
-- Create tables
CREATE TABLE contacts (
    contact_id SERIAL PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL
);

CREATE TABLE category (
    category_id SERIAL PRIMARY KEY,
    category VARCHAR(255) NOT NULL
);

CREATE TABLE subcategory (
    subcategory_id SERIAL PRIMARY KEY,
    subcategory VARCHAR(255) NOT NULL
);

CREATE TABLE campaign (
    cf_id SERIAL PRIMARY KEY,
    contact_id INTEGER NOT NULL REFERENCES contacts(contact_id),
    company_name VARCHAR(255) NOT NULL,
    description TEXT,
    goal DECIMAL(10,2) NOT NULL,
    pledged DECIMAL(10,2) NOT NULL,
    outcome VARCHAR(255),
    backers_count INTEGER NOT NULL,
    country VARCHAR(255) NOT NULL,
    currency VARCHAR(3) NOT NULL,
    launch_date DATE NOT NULL,
    end_date DATE NOT NULL,
    staff_pick BOOLEAN,
    spotlight BOOLEAN,
    category_id INTEGER NOT NULL REFERENCES category(category_id),
    subcategory_id INTEGER NOT NULL REFERENCES subcategory(subcategory_id)
);

-- Import data from CSV files
COPY contacts(contact_id, full_name, email) FROM 'contacts.csv' DELIMITER ',' CSV HEADER;
COPY category(category_id, category) FROM 'category.csv' DELIMITER ',' CSV HEADER;
COPY subcategory(subcategory_id, subcategory) FROM 'subcategory.csv' DELIMITER ',' CSV HEADER;
COPY campaign(cf_id, contact_id, company_name, description, goal, pledged, outcome, backers_count, country, currency, launch_date, end_date, staff_pick, spotlight, category_id, subcategory_id) FROM 'campaign.csv' DELIMITER ',' CSV HEADER;

-- Verify data in tables
SELECT * FROM contacts;
SELECT * FROM category;
SELECT * FROM subcategory;
SELECT * FROM campaign;

