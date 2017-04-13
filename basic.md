You're building an application that requires user login. Once logged in the user has a bunch of profile information and preference settings available to them. They will need to be able set their birthday, gender, phone number and location (city, state, country). They should be able to provide text to tell about themselves. They also should be able to enable and disable visibility of their birthday, gender, phone number and location.

user
{
  birthday: date
  gender: char
  phone number: string
  location: {
    city: string,
    state: string,
    country: string
  }
  about: String
  visibilitySettings: {
    birthdayIsVisible : boolean,
     genderIsVisible : boolean,
     phoneNumberIsVisible : boolean,
     locationIsVisible: boolean
  }
}

validation
{
  birthday: Should be reasonable human age (between 13-110 yrs old)
  gender: Should be m, f, o, mtf, ftm, nb
  phone number: Regex, all numbers, like this format (xxx) xxx-xxxx
  location: {
    city: ASCII a-z/A-Z (accents and etc)
    state: ASCII a-z/A-Z
    country: a-z/A-Z
  }
  about: String
  visibilitySettings: {
    birthdayIsVisible : boolean (y/n)
     genderIsVisible : boolean,
     phoneNumberIsVisible : boolean,
     locationIsVisible: boolean
  }
}
