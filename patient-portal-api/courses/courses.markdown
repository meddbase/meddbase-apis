---
layout: page
title: Courses
nav_order: 39
parent: Patient Portal API
---

# Courses

This section provides methods for working with courses.

A course is a pre-paid bundle of service credits. A patient buys a course once. Then the patient uses the credits to book appointments and other services, and does not pay for each one separately.

The word "course" has two meanings in this section:

- A **catalogue course** is a course that the chamber sells. It has a name, a price and a list of credits. [GetCourses](../courses/getcourses) and [GetCourse](../courses/getcourse) return catalogue courses.
- A **patient course** is one purchase of a catalogue course by one patient. It has its own dates, status and balances. [Purchase](../courses/purchase) creates a patient course. [GetPatientCourses](../courses/getpatientcourses) and [GetPatientCourse](../courses/getpatientcourse) return patient courses.

A catalogue course and a patient course have different keys. Do not mix them up:

- Use the key of a catalogue course in the `course` parameter.
- Use the key of a patient course in the `patient-course` parameter.

The chamber must have courses enabled. If courses are not enabled, each method in this section returns an error.

## Login

[GetCourses](../courses/getcourses) and [GetCourse](../courses/getcourse) can be called without login. In that case the client must provide the `payer-type` parameter, and it must be a charge-band sign-up code (see [Anonymous Appointment Search](../anonymous-appointment-search/anonymous-appointment-search)).

All other methods in this section need the client to provide the ASP.NET_SessionId key in a cookie (see [Login](../authentication/login)).

Courses are for patients. A manager (a referral portal user) cannot use the methods in this section when logged in. The patient must have the rights to view the patient overview and to book appointments.

## Keys and dates

- Keys are opaque strings. Send a key back to the server exactly as you received it.
- A date without a time is a string in the format `yyyy-MM-dd`.
- If an optional field has no value, the server does not send it.

## Credit allowances

A course gives credits by rules. The API shows each rule as a credit allowance. There are six types of credit allowance. See [CreditAllowanceType](../objects-and-data-types/creditallowancetype).

- A catalogue course shows what the course gives ([CreditAllowanceData](../objects-and-data-types/creditallowancedata)). It has no balances.
- A patient course shows what the patient has used and what is left ([CourseAllowanceData](../objects-and-data-types/courseallowancedata)).

## Booking under a course

A patient can book an appointment under a patient course. To do this, send the key of the patient course in the `patient-course` parameter of the appointment methods.

- The course decides the payer and the prices. The `payer-type` parameter is not used.
- The patient course must belong to the logged in patient.
- The patient course must be active, and the appointment must be inside the dates of the course.
- A patient course cannot be used together with a referral or a recall.
- The `patient-course` parameter is not available in the anonymous methods.

The methods that accept `patient-course` are [GetAppointmentTypes](../appointments/getappointmenttypes), [GetServiceTypes](../appointments/getservicetypes), [GetServices](../appointments/getservices), [GetSites](../appointments/getsites), [GetClinicians](../appointments/getclinicians), [GetProposedAppointments](../appointments/getproposedappointments), [GetProposedTimeSlots](../appointments/getproposedtimeslots), [BookProposedAppointment](../appointments/bookproposedappointment) and [BookProposedTimeSlot](../appointments/bookproposedtimeslot).
